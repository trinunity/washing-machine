import { AbsoluteFill, Sequence, Video, staticFile } from "remotion";
import { motion } from "framer-motion";

export const WashingMachineVideo = () => {
  return (
    <AbsoluteFill className="bg-black flex items-center justify-center">
      <div className="relative w-48 h-48 bg-gray-800 rounded-lg p-4 flex flex-col items-center justify-center">
        {/* Display Screen */}
        <motion.div
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ duration: 1 }}
          className="w-32 h-16 bg-gray-900 rounded-md flex items-center justify-center text-green-400 font-bold"
        >
          Ready
        </motion.div>

        {/* Suds and Water Animation */}
        <Sequence from={30} durationInFrames={60}>
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ duration: 1 }}
            className="absolute top-10 w-32 h-16 bg-blue-400 opacity-70 rounded-md"
          />
          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ duration: 1.5 }}
            className="absolute top-10 w-32 h-16 bg-white opacity-50 rounded-md"
          />
        </Sequence>
      </div>
    </AbsoluteFill>
  );
};
