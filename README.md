# AlgoBooker System

A decentralized hotel booking system built on the Algorand blockchain. This application allows users to book hotel rooms using ALGO tokens, with bookings stored as smart contract states on the Algorand blockchain.


## Features

- 🏨 Browse available hotel rooms
- 📅 Make room reservations using Algorand blockchain
- 💰 Pay with ALGO tokens
- 🎫 Manage bookings (view, cancel)
- 👛 Integration with MyAlgo wallet
- 🔒 Secure smart contract implementation
- 📱 Responsive design for all devices

## Technology Stack

- **Smart Contract**: PyTeal/Python
- **Backend**: Flask/Python
- **Frontend**: React/TypeScript
- **Blockchain**: Algorand
- **Styling**: TailwindCSS
- **Wallet**: MyAlgo Connect

## Prerequisites

- Node.js >= 14.0.0
- Python >= 3.8
- Algorand TestNet account with ALGO tokens
- MyAlgo wallet browser extension

## Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/algorand-hotel-booking.git
cd algorand-hotel-booking
```

2. Install backend dependencies
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Install frontend dependencies
```bash
cd frontend
npm install
```

4. Set up environment variables:

Create `.env` file in the backend directory:
```env
ALGORAND_APP_ID=your_app_id
ALGORAND_NODE_URL=https://testnet-api.algoexplorer.io
ALGORAND_TOKEN=your_token
HOTEL_OWNER_ADDRESS=your_hotel_owner_address
HOTEL_OWNER_PRIVATE_KEY=your_private_key
```

Create `.env` file in the frontend directory:
```env
REACT_APP_ALGORAND_APP_ID=your_app_id
REACT_APP_API_URL=http://localhost:5000
```

## Smart Contract Deployment

1. Compile the smart contract:
```bash
cd backend
python smart_contract.py
```

2. Deploy using the Algorand deployment script:
```bash
python deploy_contract.py
```

3. Update the APP_ID in your environment variables with the deployed contract ID.

## Running the Application

1. Start the backend server:
```bash
cd backend
python app.py
```

2. Start the frontend development server:
```bash
cd frontend
npm start
```

3. Access the application at `http://localhost:3000`

## Smart Contract Architecture

The smart contract implements the following operations:
- `initialize`: Set up hotel configuration
- `book_room`: Process room booking
- `cancel_booking`: Cancel existing booking
- `check_in`: Process guest check-in
- `check_out`: Process guest check-out

## API Endpoints

- POST `/api/initialize` - Initialize hotel configuration
- POST `/api/book-room` - Book a room
- POST `/api/cancel-booking` - Cancel a booking
- GET `/api/rooms` - Get available rooms
- GET `/api/bookings` - Get user bookings

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Testing

### Smart Contract Tests
```bash
cd backend/tests
python -m pytest test_smart_contract.py
```

### Frontend Tests
```bash
cd frontend
npm test
```

## Security Considerations

- Always use TestNet for development and testing
- Never share private keys or sensitive information
- Implement proper input validation
- Use atomic transactions where possible
- Implement rate limiting on API endpoints
- Follow Algorand best practices for smart contract security

## Project Structure
```
algorand-hotel-booking/
├── backend/
│   ├── smart_contract.py
│   ├── app.py
│   ├── requirements.txt
│   └── tests/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── utils/
│   │   └── App.tsx
│   ├── package.json
│   └── tsconfig.json
└── README.md
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Algorand Developer Documentation
- PyTeal Documentation
- React Documentation
- TailwindCSS Team


## Troubleshooting

### Common Issues

1. **MyAlgo Wallet Connection Issues**
   - Ensure MyAlgo wallet extension is installed
   - Check if you're on TestNet
   - Verify sufficient ALGO balance

2. **Smart Contract Deployment Failures**
   - Verify correct node URL
   - Check account has sufficient balance
   - Ensure correct permissions

3. **Transaction Errors**
   - Check transaction parameters
   - Verify correct app ID
   - Ensure sufficient balance for fees

## Roadmap

- [ ] Add support for multiple hotels
- [ ] Implement reward system
- [ ] Add review system
- [ ] Support for multiple payment tokens
- [ ] Enhanced booking management features
- [ ] Mobile app development

